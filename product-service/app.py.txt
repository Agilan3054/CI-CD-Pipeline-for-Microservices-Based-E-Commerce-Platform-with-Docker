from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/products', methods=['GET'])
def get_products():
    return jsonify({"products": ["Laptop", "Smartphone", "Tablet"]})

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5002)
